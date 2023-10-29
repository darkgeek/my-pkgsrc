# $NetBSD$

DISTNAME=	nomad-1.7.0
GITHUB_PROJECT=	nomad
GITHUB_TAG=	v${PKGVERSION_NOREV}
CATEGORIES=	sysutils
MASTER_SITES=	${MASTER_SITE_GITHUB:=darkgeek/}

MAINTAINER=	cirnatdan@NetBSD.org
HOMEPAGE=	https://github.com/darkgeek/nomad/
COMMENT=	Workload orchestrator that can deploy a mix of applications
LICENSE=	mpl-2.0

GO_DIST_BASE=	${GITHUB_PROJECT}-${PKGVERSION_NOREV}
GO_SRCPATH=	github.com/darkgeek/nomad/


do-install:
	${INSTALL_PROGRAM} ${WRKDIR}/.gopath/bin/nomad ${DESTDIR}${PREFIX}/bin

.include "go-modules.mk"
.include "../../lang/go/go-module.mk"

GOVERSSUFFIX=   121
GO_BUILD_PATTERN:= -tags="ui,release" ${GO_BUILD_PATTERN}

.include "../../mk/bsd.pkg.mk"